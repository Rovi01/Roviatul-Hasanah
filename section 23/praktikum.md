import 'package:bloc/bloc.dart';
import 'package:equatable/equatable.dart';

part 'size_event.dart';
part 'size_state.dart';

class SizeBloc extends Bloc<SizeEvent, SizeState> {
  SizeBloc() : super(SizeState(isBig: false)) {
    // bool isBig = false;
    // on<SizeEvent>(
    //   (event, emit) {
    //     if (event is ChangeSize) {
    //       // print('${!event.isBig}');
    //       bool newBig = isBig = !isBig;
    //       emit(SizeState(isBig: isBig));
    //       print('$isBig');
    //     }
    //   },
    // );
    on<SizeEvent>(
      (event, emit) {
        if (event is ChangeSize) {
          // print('${!event.isBig}');
          bool newBig = state.isBig = event.isBig;
          bool newBigss = !newBig;
          emit(SizeState(isBig: newBigss));
          print('$newBigss');
        }
      },
    );
  }
}

part of 'size_bloc.dart';

abstract class SizeEvent extends Equatable {
  const SizeEvent();

  @override
  List<Object> get props => [];
}

class ChangeSize extends SizeEvent {
  bool isBig;
  ChangeSize({required this.isBig});
  @override
  List<Object> get props => [isBig];
}

// ignore_for_file: public_member_api_docs, sort_constructors_first
part of 'size_bloc.dart';

class SizeState extends Equatable {
  bool isBig;
  SizeState({required this.isBig});

  @override
  List<Object> get props => [isBig];
}
