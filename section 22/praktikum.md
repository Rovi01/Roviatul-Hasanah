import 'package:bloc/bloc.dart';
import 'package:equatable/equatable.dart';
import 'package:state_management/models/m_contacts.dart';

part 'contact_event.dart';
part 'contact_state.dart';

class ContactBloc extends Bloc<ContactEvent, ContactState> {
  ContactBloc() : super(ContactLoading()) {
    on<LoadContact>((event, emit) async {
      await Future<void>.delayed(const Duration(seconds: 2));
      emit(
        ContactLoaded(
          items: const [ContactModel(name: 'Rayhan', phone: '082222213123')],
        ),
      );
    });
    on<AddContact>(
      (event, emit) {
        final state = this.state;
        if (state is ContactLoaded) {
          emit(
              ContactLoaded(items: List.from(state.items)..add(event.contact)));
        }
      },
    );
    on<RemoveContact>(
      (event, emit) {
        if (state is ContactLoaded) {
          final state = this.state as ContactLoaded;
          emit(ContactLoaded(
              items: List.from(state.items)..remove(event.contact)));
        }
      },
    );
  }
}

// ignore_for_file: public_member_api_docs, sort_constructors_first
part of 'contact_bloc.dart';

abstract class ContactEvent extends Equatable {
  const ContactEvent();

  @override
  List<Object> get props => [];
}

class LoadContact extends ContactEvent {
  List<ContactModel> items;
  LoadContact({this.items = const <ContactModel>[]});
  @override
  List<Object> get props => [items];
}

class AddContact extends ContactEvent {
  ContactModel contact;
  AddContact({
    required this.contact,
  });

  @override
  List<Object> get props => [contact];
}

class RemoveContact extends ContactEvent {
  final ContactModel contact;
  const RemoveContact({
    required this.contact,
  });
}


// class InitializeContactEvent extends ContactEvent {}

// class AddContact extends ContactEvent {
//   ContactModel contact;

//   AddContact({
//     required this.contact,
//   });
// }

// class RemoveContact extends ContactEvent {}

// ignore_for_file: public_member_api_docs, sort_constructors_first
part of 'contact_bloc.dart';

abstract class ContactState extends Equatable {
  const ContactState();

  @override
  List<Object> get props => [];
}

class ContactLoading extends ContactState {}

class ContactLoaded extends ContactState {
  List<ContactModel> items;

  ContactLoaded({this.items = const <ContactModel>[]});
  @override
  List<Object> get props => [items];
}